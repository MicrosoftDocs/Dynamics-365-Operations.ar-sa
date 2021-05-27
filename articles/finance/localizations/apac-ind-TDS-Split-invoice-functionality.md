---
title: وظيفة تقسيم الفاتورة
description: يصف هذا الموضوع الإعداد والوظيفة الخاصين بتقسيم الفواتير حسب عنوان التسليم ورقم حساب الضريبة (TAN).
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 7dddbb9f69a9735c2a03d2b23928f5cb92d4e0fd
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023003"
---
# <a name="split-invoice-functionality"></a><span data-ttu-id="602a6-103">وظيفة تقسيم الفاتورة</span><span class="sxs-lookup"><span data-stu-id="602a6-103">Split invoice functionality</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="602a6-104">يصف هذا الموضوع الإعداد والوظيفة الخاصين بتقسيم الفواتير حسب عنوان التسليم ورقم حساب الضريبة (TAN).</span><span class="sxs-lookup"><span data-stu-id="602a6-104">This topic describes the setup and functionality for splitting invoices by delivery address and tax account number (TAN).</span></span>

<span data-ttu-id="602a6-105">في الصفحة **محددات الحسابات الدائنة**، على علامة التبويب **عام**، حدد **إيصال استلام المنتج** أو خانة الاختيار **الفاتورة** لترحيل وتقسيم إيصال استلام منتج أو فاتورة تحتوي على عناوين تسليم مختلفة وأرقام TAN على الصفحة **أمر الشراء**.</span><span class="sxs-lookup"><span data-stu-id="602a6-105">On the **Accounts payable parameters** page, on the **General** tab, select the **Product receipt** or **Invoice** checkbox to post and split a product receipt or invoice that has different delivery addresses and TANs on the **Purchase order** page.</span></span> <span data-ttu-id="602a6-106">يتم عندئذ تقسيم الفاتورة التي تم ترحيلها حسب عنوان التسليم وTAN.</span><span class="sxs-lookup"><span data-stu-id="602a6-106">The posted invoice will then be split by delivery address and TAN.</span></span>

<span data-ttu-id="602a6-107">في علامة التبويب **تحديث ملخص**، على علامة التبويب السريعة **مقسم استنادًا إلى**، في الصف **معلومات التسليم‬**، قم بتعببن الخيار **تأكيد** أو **قائمة الانتقاء** أو **إيصال التعبئة** أو **فاتورة** إلى **نعم** لترحيل وتقسيم التأكيد أو قائمة الانتقاء أو إيصال التعبئة أو الفاتورة حيث يتم تحديد عناوين التسليم مختلفة ويتم تحديد أرقام TAN لبنود فواتير مختلفة على الصفحة **أمر المبيعات**:</span><span class="sxs-lookup"><span data-stu-id="602a6-107">On the **Summary update** tab, on the **Split based on** FastTab, in the **Delivery information** row, set the **Confirmation**, **Picking list**, **Packing slip**, or **Invoice** option to **Yes** to post and split a confirmation, picking list, packing slip, or invoice where different delivery addresses and TANs are defined for different invoice lines on the **Sales order** page.</span></span> <span data-ttu-id="602a6-108">يتم تقسيم الفاتورة أولاً حسب عنوان التسليم ثم حسب TAN.</span><span class="sxs-lookup"><span data-stu-id="602a6-108">The invoice will be split first by delivery address and then by TAN.</span></span>

> [!IMPORTANT]
> - <span data-ttu-id="602a6-109">إذا لم يتم تعيين أية خيارات لـ **معلومات التسليم** إلى **نعم**، فإنه سيتم ترحيل الفاتورة كفاتورة واحدة.</span><span class="sxs-lookup"><span data-stu-id="602a6-109">If no options for **Delivery information** are set to **Yes**, the invoice will be posted as a single invoice.</span></span> <span data-ttu-id="602a6-110">لن يحدث أي تقسيم للفاتورة.</span><span class="sxs-lookup"><span data-stu-id="602a6-110">No invoice splitting will occur.</span></span>
> - <span data-ttu-id="602a6-111">لتقسيم إيصال التعبئة وترحيله حيث تشتمل بنود الفاتورة على عناوين تسليم وأرقام TAN مختلفة، فإنه يجب أن تقوم بتعيين الخيار **إيصال التعبئة** لـ **معلومات التسليم** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="602a6-111">To split and post a packing slip where the invoice lines have different delivery addresses and TANs, you must set the **Packing slip** option for **Delivery information** to **Yes**.</span></span>
> - <span data-ttu-id="602a6-112">لتقسيم فاتورة وترحيلها حيث تشتمل بنود الفاتورة على عناوين تسليم وأرقام TAN مختلفة، ويجب أن تقوم بتعيين الخيار **الفاتورة** لـ **معلومات التسليم** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="602a6-112">To split and post an invoice where the invoice lines have different delivery addresses and TANs, you must set the **Invoice** option for **Delivery information** to **Yes**.</span></span>
> - <span data-ttu-id="602a6-113">لترحيل فاتورة حيث تشتمل بنود الفاتورة على عناوين تسليم ولكن برقم TAN نفسه، فإنه يجب أن تقوم بتعيين الخيار **الفاتورة** لـ **معلومات التسليم** إلى **لا**.</span><span class="sxs-lookup"><span data-stu-id="602a6-113">To post an invoice where the invoice lines have different delivery addresses but the same TAN, set the **Invoice** option for **Delivery information** to **No**.</span></span> <span data-ttu-id="602a6-114">يتم تقسيم الفاتورة حسب عنوان التسليم.</span><span class="sxs-lookup"><span data-stu-id="602a6-114">The invoice will be split by delivery address.</span></span>

## <a name="example"></a><span data-ttu-id="602a6-115">مثال</span><span class="sxs-lookup"><span data-stu-id="602a6-115">Example</span></span>

<span data-ttu-id="602a6-116">في هذا المثال، يتم تعيين الخيار **الفاتورة** الخاص بـ **معلومات التسليم** إلى **نعم** في علامة التبويب **تحديث الملخص** لصفحة **معلمات الحسابات الدائنة**.</span><span class="sxs-lookup"><span data-stu-id="602a6-116">In this example, the **Invoice** option for **Delivery information** is set to **Yes** on the **Summary update** tab of the **Accounts payable parameters** page.</span></span> <span data-ttu-id="602a6-117">يتم ترحيل فاتورة الشراء التي تحتوي على الإعداد التالي لعناوين التسليم وأرقام TAN على البنود:</span><span class="sxs-lookup"><span data-stu-id="602a6-117">A purchase invoice is posted that has the following setup for delivery addresses and TANs on the lines:</span></span>

- <span data-ttu-id="602a6-118">**بند الصنف 1:** عنوان التسليم 1، TAN-ABCD12345A</span><span class="sxs-lookup"><span data-stu-id="602a6-118">**Item line 1:** Delivery address 1, TAN-ABCD12345A</span></span>
- <span data-ttu-id="602a6-119">**بند الصنف 2:** عنوان التسليم 1، TAN-ABCD12345A</span><span class="sxs-lookup"><span data-stu-id="602a6-119">**Item line 2:** Delivery address 1, TAN-ABCD12345A</span></span>
- <span data-ttu-id="602a6-120">**بند الصنف 3:** عنوان التسليم 2، TAN-ABCE12345B</span><span class="sxs-lookup"><span data-stu-id="602a6-120">**Item line 3:** Delivery address 2, TAN-ABCE12345B</span></span>
- <span data-ttu-id="602a6-121">**بند الصنف 4:** عنوان التسليم 3، TAN-ABCD12345A</span><span class="sxs-lookup"><span data-stu-id="602a6-121">**Item line 4:** Delivery address 3, TAN-ABCD12345A</span></span>

<span data-ttu-id="602a6-122">في هذه الحالة، يتم تقسيم الفاتورة الأصلية إلى فاتورتين ويتم ترحيلها بالطريقة التالية:</span><span class="sxs-lookup"><span data-stu-id="602a6-122">In this case, the original invoice is split into two invoices and posted in the following way:</span></span>

- <span data-ttu-id="602a6-123">يتم ترحيل الفاتورة 1 لبند الصنف 1 وبند الصنف 2، لأن كلا البندين يشتملان على عنوان التسليم نفسه ورقم TAN نفسه.</span><span class="sxs-lookup"><span data-stu-id="602a6-123">Invoice 1 is posted for item line 1 and item line 2, because both lines have the same delivery address and TAN.</span></span>
- <span data-ttu-id="602a6-124">يتم ترحيل الفاتورة 2 لبند الصنف 3.</span><span class="sxs-lookup"><span data-stu-id="602a6-124">Invoice 2 is posted for item line 3.</span></span>
- <span data-ttu-id="602a6-125">يتم ترحيل الفاتورة 3 لبند الصنف 4.</span><span class="sxs-lookup"><span data-stu-id="602a6-125">Invoice 3 is posted for item line 4.</span></span>
