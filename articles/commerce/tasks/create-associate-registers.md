---
title: " إنشاء وربط سجلات"
description: يوضح هذا الإجراء كيفية إنشاء سجل نقطة البيع.
author: rubencdelgado
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailTerminalTable
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: af9743f17cebb3484c3ec5b0315347c575a474bd
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5246985"
---
# <a name="create-and-associate-registers"></a><span data-ttu-id="03d37-103"> إنشاء وربط سجلات</span><span class="sxs-lookup"><span data-stu-id="03d37-103">Create and associate registers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="03d37-104">يوضح هذا الإجراء كيفية إنشاء سجل نقطة البيع.</span><span class="sxs-lookup"><span data-stu-id="03d37-104">This procedure demonstrates how to create a point of sale (POS) register.</span></span> <span data-ttu-id="03d37-105">يستخدم هذا الإجراء شركة بيانات العرض التوضيحي USRT.</span><span class="sxs-lookup"><span data-stu-id="03d37-105">This procedure uses the demo data company USRT.</span></span>

1. <span data-ttu-id="03d37-106">انتقل إلى البيع بالتجزئة والتجارة > إعداد القناة > إعداد نقطة البيع > السجلات.</span><span class="sxs-lookup"><span data-stu-id="03d37-106">Go to Retail and Commerce > Channel setup > POS setup > Registers.</span></span>
2. <span data-ttu-id="03d37-107">انقر فوق جديد.</span><span class="sxs-lookup"><span data-stu-id="03d37-107">Click New.</span></span>
3. <span data-ttu-id="03d37-108">في الحقل "رقم السجل" اكتب معرف السجل الجديد.</span><span class="sxs-lookup"><span data-stu-id="03d37-108">In the Register number field, type an ID for the new register.</span></span>
    * <span data-ttu-id="03d37-109">يتضمن "معرف السجل" عادةً أكوادًا قد تساعد على تعيين السجل إلى المتجر الذي ينتمي إليه والموقع داخل المخزن.</span><span class="sxs-lookup"><span data-stu-id="03d37-109">The register ID typically includes codes that help map the register to the store to which it belongs, and the location within the store.</span></span>  
4. <span data-ttu-id="03d37-110">في حقل "الاسم"، اكتب اسمًا وصفيًا للسجل.</span><span class="sxs-lookup"><span data-stu-id="03d37-110">In the Name field, type a descriptive name for the register..</span></span>
5. <span data-ttu-id="03d37-111">في الحقل "رقم المتجر"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="03d37-111">In the Store number field, enter or select a value.</span></span>
6. <span data-ttu-id="03d37-112">في الحقل "ملف تعريف الأجهزة"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="03d37-112">In the Hardware profile field, enter or select a value.</span></span>
    * <span data-ttu-id="03d37-113">يتم استخدام ملفات تعريف الأجهزة لتحديد الأجهزة الطرفية التي سيتم توصيلها بالسجل، مثل درج الأوراق النقدية وطابعة الإيصالات.</span><span class="sxs-lookup"><span data-stu-id="03d37-113">Hardware profiles are used to specify the peripherals that will be connected to the register, such as cash drawer and receipt printer.</span></span>  
7. <span data-ttu-id="03d37-114">في حقل "ملف التعريف المرئي‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="03d37-114">In the Visual profile field, enter or select a value.</span></span>
    * <span data-ttu-id="03d37-115">يتم استخدام ملفات التعريف المرئية لتحديد الصور المستخدمة في خلفية نقطة البيع وصفحة تسجيل الدخول بالإضافة إلى نُسق نقطة البيع.</span><span class="sxs-lookup"><span data-stu-id="03d37-115">Visual profiles are used to specify the images used in the POS background and login page as well as themes for the POS.</span></span>  
8. <span data-ttu-id="03d37-116">في الحقل "رقم تسجيل نقطة بيع EFT"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="03d37-116">In the EFT POS register number field, type a value.</span></span>
    * <span data-ttu-id="03d37-117">يتم استخدام "رقم تسجيل نقطة بيع EFT" لإعلام معالج الدفع بمحطة الدفع الطرفية التي تُرسل طلبات التفويض.</span><span class="sxs-lookup"><span data-stu-id="03d37-117">The EFT POS register number is used to inform the payment processor which payment terminal is sending authorization requests.</span></span> <span data-ttu-id="03d37-118">غالبًا ما تسمى هذه القيمة "معرف المحطة الطرفية" أو "TID".</span><span class="sxs-lookup"><span data-stu-id="03d37-118">This value is often called the "Terminal ID" or "TID".</span></span> <span data-ttu-id="03d37-119">يمكن العثور على TID عادةً على ملصق على جهاز الدفع.</span><span class="sxs-lookup"><span data-stu-id="03d37-119">The TID can generally be found on a sticker on the payment device.</span></span>  
9. <span data-ttu-id="03d37-120">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="03d37-120">Click Save.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]