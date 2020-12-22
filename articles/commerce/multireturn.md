---
title: إرجاع أصناف عبر عدة فواتير وأوامر مبيعات للعملاء
description: يوضح هذا الموضوع الوظيفة التي تمكّن عمليات الإرجاع عبر العديد من الفواتير وأوامر العملاء في Dynamics 365 Commerce.
author: josaw1
manager: AnnBe
ms.date: 08/27/2020
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-01-15
ms.dyn365.ops.version: 10
ms.openlocfilehash: e95f06ffaaf2d250b02a8458faa2d9e0b5ef5631
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/13/2020
ms.locfileid: "4458353"
---
# <a name="return-items-across-multiple-customer-orders-and-invoices"></a><span data-ttu-id="d7730-103">إرجاع أصناف عبر عدة فواتير وأوامر مبيعات للعملاء</span><span class="sxs-lookup"><span data-stu-id="d7730-103">Return items across multiple customer orders and invoices</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="d7730-104">يصف هذا المقال وظيفتين لتحسين عمليات إرجاع أوامر العملاء عبر عدة فواتير.</span><span class="sxs-lookup"><span data-stu-id="d7730-104">This article describes two features that optimize customer order returns over multiple invoices.</span></span> 

## <a name="enable-refunds-over-multiple-captures"></a><span data-ttu-id="d7730-105">تمكين المبالغ المستردة عبر عمليات الالتقاط المتعددة</span><span class="sxs-lookup"><span data-stu-id="d7730-105">Enable refunds over multiple captures</span></span>

<span data-ttu-id="d7730-106">تُمكن هذه الميزة العديد من المبالغ المستردة المرتبطة لنفس أمر العميل.</span><span class="sxs-lookup"><span data-stu-id="d7730-106">This feature enables multiple linked refunds against the same customer order.</span></span> 

1. <span data-ttu-id="d7730-107">انتقل إلى مساحة عمل **إدارة الميزات** وابحث عن **‏‫تمكين المبالغ المستردة عبر عمليات الالتقاط المتعددة‬**.</span><span class="sxs-lookup"><span data-stu-id="d7730-107">Go to the **Feature management** workspace and search for **Enable refunds over multiple captures**.</span></span>
2. <span data-ttu-id="d7730-108">حدد **‏‫تمكين المبالغ المستردة عبر عمليات الالتقاط المتعددة‬** ثم انقر **تمكين**.</span><span class="sxs-lookup"><span data-stu-id="d7730-108">Select **Enable refunds over multiple orders** and then click **Enable**.</span></span> 

## <a name="enable-proper-tax-calculation-for-returns-with-partial-quantity"></a><span data-ttu-id="d7730-109">تمكين الحساب المناسب للضريبة للمرتجعات التي تحتوي على كمية جزئية</span><span class="sxs-lookup"><span data-stu-id="d7730-109">Enable proper tax calculation for returns with partial quantity</span></span>

<span data-ttu-id="d7730-110">تضمن هذه الوظيفة مساواة الضرائب في النهاية لمبلغ الضريبة المحصل بالأصل وذلك عند إرجاع أمر باستخدام فواتير متعددة.</span><span class="sxs-lookup"><span data-stu-id="d7730-110">This feature ensures that when an order is returned using multiple invoices, the taxes will ultimately be equal to the tax amount originally charged.</span></span> 

1. <span data-ttu-id="d7730-111">انتقل إلى مساحة عمل **إدارة الميزات** وابحث عن **‏‫‏‫تمكين الحساب المناسب للضريبة للمرتجعات التي تحتوي على كمية جزئية‬**.</span><span class="sxs-lookup"><span data-stu-id="d7730-111">Go to the **Feature management** workspace and search for **Enable proper tax calculation for returns with partial quantity**.</span></span>
2. <span data-ttu-id="d7730-112">حدد **تمكين الحساب المناسب للضريبة للمرتجعات التي تحتوي على كمية جزئية** ثم انقر **تمكين**.</span><span class="sxs-lookup"><span data-stu-id="d7730-112">Select **Enable proper tax calculation for returns with partial quantity** and then click **Enable**.</span></span> 


## <a name="process-returns"></a><span data-ttu-id="d7730-113">معالجة المرتجعات</span><span class="sxs-lookup"><span data-stu-id="d7730-113">Process returns</span></span>

<span data-ttu-id="d7730-114">بعد تشغيل هذه الوظائف ومزامنة التغييرات مع المتاجر، بإمكان أمين الصندوق في المتجر تحديد أوامر مبيعات متعددة لعميل لمعالجة المرتجعات.</span><span class="sxs-lookup"><span data-stu-id="d7730-114">After these features are turned on and the changes are synchronized to the stores, the cashier in the store can select multiple sales orders for a customer for their return.</span></span>

<span data-ttu-id="d7730-115">عند تحديد الأوامر، تظهر قائمة بكافة المنتجات القابلة للإرجاع عبر كافة الفواتير الخاصة بالأوامر.</span><span class="sxs-lookup"><span data-stu-id="d7730-115">When the orders are selected, a list of all the returnable products across all the invoices for the orders will display.</span></span> <span data-ttu-id="d7730-116">بإمكان أمين الصندوق عندئذٍ تحديد المنتجات المطلوب إرجاعها.</span><span class="sxs-lookup"><span data-stu-id="d7730-116">The cashier can then select the products to return.</span></span> <span data-ttu-id="d7730-117">سيتم إنشاء أمر إرجاع واحد لكافة المنتجات المحددة.</span><span class="sxs-lookup"><span data-stu-id="d7730-117">A single return order will be created for all the selected products.</span></span>

<span data-ttu-id="d7730-118">في حالة إرجاع الأمر بالكامل، يكون مبلغ الضرائب المرتجع إلى العميل مساويًا لمبلغ الضريبة المحصل بالأصل.</span><span class="sxs-lookup"><span data-stu-id="d7730-118">If the order is fully returned, the amount of taxes returned to the customer will be equal to the amount of tax originally charged.</span></span>

