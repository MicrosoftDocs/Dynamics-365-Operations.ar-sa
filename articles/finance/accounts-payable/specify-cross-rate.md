---
title: تحديد سعر الصرف المتداخل
description: يقدم هذا الموضوع معلومات حول الأسعار المتداخلة في Microsoft Dynamics 365 Finance.
author: abruer
manager: AnnBe
ms.date: 05/16/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 146794557a3a6ba1801598fe6b814e209d9f5fc6
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/27/2019
ms.locfileid: "2176291"
---
# <a name="specify-the-cross-rate"></a><span data-ttu-id="a07a0-103">تحديد سعر الصرف المتداخل</span><span class="sxs-lookup"><span data-stu-id="a07a0-103">Specify the cross rate</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a07a0-104">يشرح هذا الموضوع الغرض من سعر الصرف المتداخل وكيفية تحديد سعر الصرف المتداخل عند تسوية دفع باستخدام فاتورة.</span><span class="sxs-lookup"><span data-stu-id="a07a0-104">This topic explains the purpose of a cross rate, and how to specify the cross rate when you settle a payment with an invoice.</span></span> <span data-ttu-id="a07a0-105">استخدم سعر الصرف المتداخل عند تطبيق جميع المعايير التالية:</span><span class="sxs-lookup"><span data-stu-id="a07a0-105">Use a cross rate when all of the following criteria apply:</span></span> 
-   <span data-ttu-id="a07a0-106">تسوية دفعة بفاتورة.</span><span class="sxs-lookup"><span data-stu-id="a07a0-106">You are settling a payment with an invoice.</span></span> 
-   <span data-ttu-id="a07a0-107">يستخدم كل من بند الدفع وبند الفاتورة عملات مختلفة.</span><span class="sxs-lookup"><span data-stu-id="a07a0-107">The payment line and the invoice line use different currencies.</span></span> 
-   <span data-ttu-id="a07a0-108">عمله المحاسبة ليست إحدى هاتين العملتين.</span><span class="sxs-lookup"><span data-stu-id="a07a0-108">Neither currency is the accounting currency.</span></span> 

<span data-ttu-id="a07a0-109">لا تستخدم أسعار الصرف المتداخلة لحساب تحويل عملة حركة الدفع إلى عملة محاسبة الدفع.</span><span class="sxs-lookup"><span data-stu-id="a07a0-109">The cross rate is not used to calculate the payment transaction currency translation to the payment accounting currency.</span></span> <span data-ttu-id="a07a0-110">بدلًا من ذلك، يتم استرداد أسعار الصرف من جداول أسعار الصرف لحساب قيمة مبلغ عملة حركة الدفع ومبلغ عملة محاسبة الدفع.</span><span class="sxs-lookup"><span data-stu-id="a07a0-110">Instead, the exchange rates from the exchange rate tables are retrieved to calculate the value of the payment transaction currency amount and the payment accounting currency amount.</span></span> 

<span data-ttu-id="a07a0-111">على سبيل المثال، عملة المحاسبة هي الدولار الأمريكي وعملة الفاتورة هي الدولار الكندي وعملة الدفع هي اليورو.</span><span class="sxs-lookup"><span data-stu-id="a07a0-111">For example, the accounting currency is USD, the invoice currency is CAD, and the payment currency is EUR.</span></span> <span data-ttu-id="a07a0-112">يسمح لك سعر الصرف المتداخل من إدخال سعر الصرف للتحويل مباشرةً بين اليورو والدولار الكندي، وليس من الضروري التحويل من الدولار الأمريكي.</span><span class="sxs-lookup"><span data-stu-id="a07a0-112">The cross rate lets you enter an exchange rate to translate directly between CAD and EUR, and not have to translate through USD.</span></span> <span data-ttu-id="a07a0-113">وعند تحديد فاتورة وعملية دفع أساسية، يمكن إدخال سعر الصرف المتداخل لبند الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="a07a0-113">When you select an invoice and a primary payment, you can enter a cross rate for the invoice line.</span></span> <span data-ttu-id="a07a0-114">ويكون سعر البند المتداخل هو سعر الصرف بين العملات لهذه الحركات كما هي في تاريخ التسوية.</span><span class="sxs-lookup"><span data-stu-id="a07a0-114">The cross rate is the exchange rate between the currencies for those transactions, as of the settlement date.</span></span>

1.  <span data-ttu-id="a07a0-115">انتقل إلى أحد الصفحات التالية:</span><span class="sxs-lookup"><span data-stu-id="a07a0-115">Go to one of the following pages:</span></span>
- <span data-ttu-id="a07a0-116">**الحسابات المدينة > مشترك > العملاء > كافة العملاء**</span><span class="sxs-lookup"><span data-stu-id="a07a0-116">**Accounts receivable > Common > Customers > All customers**</span></span> 
- <span data-ttu-id="a07a0-117">**الحسابات الدائنة > مشترك > المورّدون‬ > كافة الموردين**</span><span class="sxs-lookup"><span data-stu-id="a07a0-117">**Accounts payable > Common > Vendors > All vendors**</span></span> 
- <span data-ttu-id="a07a0-118">**‏‫التدبير والتوريد > مشترك > الموردون > كافة الموردين‏‫.**</span><span class="sxs-lookup"><span data-stu-id="a07a0-118">**Procurement and sourcing > Common > Vendors > All vendors**</span></span>
2.  <span data-ttu-id="a07a0-119">حدد العميل أو المورد الذي تقوم بتسوية الحركات المفتوحة الخاصة به.</span><span class="sxs-lookup"><span data-stu-id="a07a0-119">Select the customer or vendor whose open transactions you are settling.</span></span> 
3.  <span data-ttu-id="a07a0-120">بالنسبة لعميل، في صفحة قائمة **كافة العملاء**، انتقل إلى **تحصيل > تسوية الحركات المفتوحة**.</span><span class="sxs-lookup"><span data-stu-id="a07a0-120">For a customer, on the **All customers** list page, go to **Collect > Settle open transactions**.</span></span> <span data-ttu-id="a07a0-121">بالنسبة للمورد، في صفحة قائمة **كافة الموردين**، انتقل إلى **فاتورة > تسوية الحركات المفتوحة**.</span><span class="sxs-lookup"><span data-stu-id="a07a0-121">For a vendor, on the **All vendors** list page, go to **Invoice > Settle open transactions**.</span></span> 
4.  <span data-ttu-id="a07a0-122">حدد الحركة التي تعتبر عملية دفع أساسية، ثم انقر فوق زر **تمييز عملية الدفع**.</span><span class="sxs-lookup"><span data-stu-id="a07a0-122">Select the transaction that is the primary payment, and then click **Mark payment**.</span></span> <span data-ttu-id="a07a0-123">يتم تحديد خانة الاختيار الموجودة في العمود **وضع علامة**، كما يتم عرض رمز معلومات في عمود **عملية دفع أساسية** .</span><span class="sxs-lookup"><span data-stu-id="a07a0-123">The check box in the **Mark** column is selected, and an information icon is shown in the **Primary payment** column.</span></span> 
5.  <span data-ttu-id="a07a0-124">في حقل **سعر الصرف المتداخل**، ادخل سعر الصرف بين عملة الفاتورة وعملة الدفع، اعتبارًا من تاريخ التسوية.</span><span class="sxs-lookup"><span data-stu-id="a07a0-124">In the **Cross rate** field, enter the exchange rate between the invoice currency and the payment currency, as of the settlement date.</span></span> 
