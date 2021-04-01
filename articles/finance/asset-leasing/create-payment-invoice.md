---
title: إنشاء فواتير دفع
description: يشرح هذا الموضوع كيفية إنشاء فواتير عقود الإيجار الشهرية‬. يمكنك إنشاء فواتير فردية لعقود الإيجار، أو يمكنك استخدام معالجة الدُفعة لإنشاءها للعديد من عقود الإيجار.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: a8b9457b158afaa32718976a7a97f48411be0e1a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5241512"
---
# <a name="create-payment-invoices"></a><span data-ttu-id="f5775-104">إنشاء فواتير دفع</span><span class="sxs-lookup"><span data-stu-id="f5775-104">Create payment invoices</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f5775-105">يمكنك إنشاء فواتير فردية لعقود الإيجار شهرية، أو يمكنك استخدام معالجة الدُفعة لإنشاءها للعديد من عقود الإيجار.</span><span class="sxs-lookup"><span data-stu-id="f5775-105">You can create monthly invoices for individual leases, or you can use a batch process to create them for multiple leases.</span></span> <span data-ttu-id="f5775-106">يوضح الإجراء التالي كيفية إنشاء إدخال دفعات الإيجار الفردية عند تشغيل المعلمة **الدفع إلى المورد** في الصفحة **إعداد دفتر الإيجار**.</span><span class="sxs-lookup"><span data-stu-id="f5775-106">The following procedure shows how to create an individual lease payment entry when the **Pay to Vendor** parameter on the **Lease book setup** page is turned on.</span></span>

1. <span data-ttu-id="f5775-107">في الصفحة **ملخص عقد الإيجار**، حدد عقد إيجار، ثم حدد **الدفاتر \> جدول الدفع**.</span><span class="sxs-lookup"><span data-stu-id="f5775-107">On the **Lease summary** page, select a lease, and then select **Books \> Payment schedule**.</span></span>
2. <span data-ttu-id="f5775-108">حدد الدفع الذي يجب القيام به، ثم حدد **إنشاء دفتر اليومية**.</span><span class="sxs-lookup"><span data-stu-id="f5775-108">Select the payment that must be made, and then select **Create journal**.</span></span> <span data-ttu-id="f5775-109">وتظهر رسالة توضح أنه تم إنشاء دفتر يومية مقابل عملية الدفع المحددة.</span><span class="sxs-lookup"><span data-stu-id="f5775-109">You receive a message that states that a journal was created against the selected payment.</span></span>
3. <span data-ttu-id="f5775-110">حدد **دفاتر يومية الفاتورة**، ثم حدد الفاتورة التي يجب دفعها.</span><span class="sxs-lookup"><span data-stu-id="f5775-110">Select **Invoice journals**, and then select the invoice that must be paid.</span></span>
4. <span data-ttu-id="f5775-111">من علامة التبويب **البنود**، راجع إدخال دفتر اليومية قبل ترحيله إلى دفتر الأستاذ العام.</span><span class="sxs-lookup"><span data-stu-id="f5775-111">On the **Lines** tab, review the journal entry before you post it to the general ledger.</span></span>

    > [!NOTE]
    > <span data-ttu-id="f5775-112">بشكل افتراضي ، تقوم بنود فاتورة المورد التي تم إنشاؤها باستخدام ملف تعريف ترحيل المورد من الصفحة **معلمات الحسابات الدائنة**.</span><span class="sxs-lookup"><span data-stu-id="f5775-112">By default, the vendor invoice lines that are created use the vendor posting profile from the **Accounts payable parameters** page.</span></span>

5. <span data-ttu-id="f5775-113">حدد دفتر اليومية الصحيح، ثم حدد الفاتورة التي يجب دفعها.</span><span class="sxs-lookup"><span data-stu-id="f5775-113">Select the correct journal, and then select the invoice that must be paid.</span></span>

    <span data-ttu-id="f5775-114">بالنسبة لهذا المثال، يتم تشغيل المعلمة **الدفع إلى المورد** في دفتر الإيجار.</span><span class="sxs-lookup"><span data-stu-id="f5775-114">For this example, the **Pay to Vendor** parameter on the lease book is turned on.</span></span> <span data-ttu-id="f5775-115">وبالتالي، ستكون الفاتورة في دفتر يومية الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="f5775-115">Therefore, the invoice will be in the invoice journal.</span></span> <span data-ttu-id="f5775-116">يعرض القسم **نظرة عامة** ملخصًا لإدخال دفتر اليومية، ويعرض القسم **البنود** تفاصيل بنود دفتر اليومية الفعلية.</span><span class="sxs-lookup"><span data-stu-id="f5775-116">The **Overview** section shows a summary of the journal entry, and the **Lines** section shows details of the actual journal lines.</span></span>

    > [!NOTE]
    > <span data-ttu-id="f5775-117">في حالة إيقاف تشغيل المعلمة **الدفع إلى المورد**، فإنه سيتم إدراج إدخالات دفتر يومية المدفوعات في الصفحة **تأجير الأصول** لدفتر الإيجار، وسيقوم النظام بإنشاء إدخال تأجير الأصل بدلاً من الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="f5775-117">If the **Pay to Vendor** parameter is turned off, payment journal entries will be listed on the **Asset leasing** page for the lease book, and the system will create an asset leasing entry instead of an invoice.</span></span> <span data-ttu-id="f5775-118">سيتم ترحيل إدخال دفعات الإيجار إلى اسم دفتر اليومية المحدد في الحقل **دفتر يومية عقد الإيجار شهريًا**.</span><span class="sxs-lookup"><span data-stu-id="f5775-118">The lease payment entry will be posted to the journal name that is specified in the **Monthly lease journal** field.</span></span>

6. <span data-ttu-id="f5775-119">بعد ترحيل الحركة، فإنه يمكنك عرض معلومات الحركة وقيمة الحمل الخاصة بالتزامات الإيجار عن طريق تحديد **حركات الالتزام** في دفتر الإيجار.</span><span class="sxs-lookup"><span data-stu-id="f5775-119">After the transaction is posted, you can view the transaction information and the carrying value of the lease liability by selecting **Liability transactions** in the lease book.</span></span>

    <span data-ttu-id="f5775-120">في جدول الدفع، سيتم تحديد خانة الاختيار **دفتر اليومية مُرحل**، وسيعرض البند رقم دفتر يومية الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="f5775-120">In the payment schedule, the **Journal posted** check box will be selected, and the line will show the invoice journal number.</span></span> <span data-ttu-id="f5775-121">بعد إنشاء دفتر يومية المدفوعات وإدخال لدفتر اليومية ذلك، فإنه يجب عليك إلغاء الإدخال قبل إعادة إنشائه.</span><span class="sxs-lookup"><span data-stu-id="f5775-121">After a payment journal and an entry for that journal have been created, you must reverse the entry before it can be re-created.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]